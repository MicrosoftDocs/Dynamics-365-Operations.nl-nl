---
title: Callcenterfunctionaliteit
description: Dit onderwerp bevat een overzicht van de verkoopfunctionaliteit voor callcenters in Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 52b3e2e78a03ac67507ee65a03e0884e5ed44678
ms.openlocfilehash: 75dc09ffc84ef8ec48f50ea410974c99aabc212e
ms.contentlocale: nl-nl
ms.lasthandoff: 11/14/2017

---

# <a name="call-center-functionality"></a><span data-ttu-id="a36ac-103">Callcenterfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="a36ac-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a36ac-104">Dit artikel bevat een overzicht van de verkoopfunctionaliteit voor callcenters in Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="a36ac-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="a36ac-105">Dynamics 365 for Retail ondersteunt ook callcenters als type detailhandelkanaal.</span><span class="sxs-lookup"><span data-stu-id="a36ac-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="a36ac-106">In een callcenter nemen werknemers telefonische orders aan van klanten en maken ze verkooporders.</span><span class="sxs-lookup"><span data-stu-id="a36ac-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="a36ac-107">De callcenterfunctie omvat functies die zijn ontworpen om het gemakkelijker te maken om telefoonorders aan te nemen en klantenservice te bieden door het orderverwerkingsproces heen.</span><span class="sxs-lookup"><span data-stu-id="a36ac-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="a36ac-108">Bijvoorbeeld: medewerkers van callcenters kunnen betalingsgegevens rechtstreeks invoeren in de verkooporder en een gedetailleerd overzicht van de toeslagen en betalingen bekijken voordat ze de order indienen.</span><span class="sxs-lookup"><span data-stu-id="a36ac-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="a36ac-109">Werknemers hebben ook opties om prijzen te regelen en kunnen uiteenlopende gegevens bekijken over klanten, producten en prijzen van de **verkooporderpagina**.</span><span class="sxs-lookup"><span data-stu-id="a36ac-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="a36ac-110">Daarnaast hebben callcenters ook verbeterde functionaliteit voor het bijhouden van klanthistorie en orderstatus.</span><span class="sxs-lookup"><span data-stu-id="a36ac-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="a36ac-111">Elk call center kan eigen gebruikers, betalingsmethoden, prijsgroepen, financiële dimensies en leveringsmethoden hebben.</span><span class="sxs-lookup"><span data-stu-id="a36ac-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="a36ac-112">U kunt deze opties configureren wanneer u het call center maakt.</span><span class="sxs-lookup"><span data-stu-id="a36ac-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="a36ac-113">Bovendien, kunt u de pagina **Callcenter** gebruiken om de volgende groepen functies in te schakelen of uit te schakelen die uniek voor callcenters:</span><span class="sxs-lookup"><span data-stu-id="a36ac-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="a36ac-114">**Ordervoltooiing**: deze groep bevat functies die aan betalingen en ordervoltooiing in de **Verkooporder** zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="a36ac-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="a36ac-115">**Geleide verkoop:** deze groep bevat functies die aan broncodes, scripts en catalogusaanvragen worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="a36ac-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="a36ac-116">Wanneer u deze functies in de instellingen van het call center inschakelt, worden ze beschikbaar in de **Verkooporder** pagina voor gebruikers die aan het call center worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="a36ac-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="a36ac-117">De meeste van deze functies vereisen aanvullende instellingen voordat ze gebruikt kunnen worden.</span><span class="sxs-lookup"><span data-stu-id="a36ac-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="a36ac-118">Voordat gebruikers de orders van het callcenter kunnen maken, moet u die gebruikers toevoegen aan het callcenter als gebruikers van het callcenter.</span><span class="sxs-lookup"><span data-stu-id="a36ac-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="a36ac-119">Deze stap schakelt het callcenterkanaal-specifieke configuratie en de functionaliteit in.</span><span class="sxs-lookup"><span data-stu-id="a36ac-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="a36ac-120">Hieronder staan enkele voorbeelden van de funktionaliteit die beschikbaar wordt:</span><span class="sxs-lookup"><span data-stu-id="a36ac-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="a36ac-121">Geleide verkoop biedt configuratieopties voor telesalesscripts en productafbeeldingen om verkoopbedienden te helpen en te begeleiden terwijl deze orders aannemen.</span><span class="sxs-lookup"><span data-stu-id="a36ac-121">Guided selling provides configuration options for tele-sales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="a36ac-122">De orders kunnen niet worden voltooid totdat de verkoopbedienden minimaal één betalingsmethode hebben vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="a36ac-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="a36ac-123">Upsell en cross-sell regels kunnen worden geconfigureerd om verkoopbedienden aan te moedigen om specifieke producten naar de klant te promoten.</span><span class="sxs-lookup"><span data-stu-id="a36ac-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="a36ac-124">Verkoopbedienden kunnen de broncode voor de catalogus waaruit een klant bestelt lezen.</span><span class="sxs-lookup"><span data-stu-id="a36ac-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="a36ac-125">Verkoopbedienden kunnen de coupons van een detailhandelaar aan de order toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a36ac-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="a36ac-126">Verkoopbedienden kunnen continuïteitsprogramma's verkopen.</span><span class="sxs-lookup"><span data-stu-id="a36ac-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="a36ac-127">De orders kunnen worden handmatig geblokkeerd worden, om aan te geven dat het verder onderzoek is vereist voordat de order kan worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="a36ac-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





