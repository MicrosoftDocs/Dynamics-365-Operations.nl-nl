---
title: Callcenterfunctionaliteit
description: Dit onderwerp bevat een overzicht van de verkoopfunctionaliteit voor callcenters in Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
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
ms.sourcegitcommit: 6e4f89d86b64e0c8c76c15d3c2c1c00af353e9ca
ms.openlocfilehash: e76b29cf6312959ee84c251d582310ce4822945f
ms.contentlocale: nl-nl
ms.lasthandoff: 05/17/2018

---

# <a name="call-center"></a><span data-ttu-id="4d78a-103">Callcenter</span><span class="sxs-lookup"><span data-stu-id="4d78a-103">Call center</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="4d78a-104">In Dynamics 365 for Retail is een callcenter een type detailhandelafzetkanaal dat kan worden gedefinieerd in de toepassing.</span><span class="sxs-lookup"><span data-stu-id="4d78a-104">In Dynamics 365 for Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="4d78a-105">Als u een specifiek kanaal definieert voor uw callcenterentiteiten, kan het systeem specifieke gegevensstandaardwaarden en standaardwaarden voor orderverwerking koppelen aan verkooporders die zijn gemaakt door een gebruiker of het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="4d78a-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="4d78a-106">Callcenterfuncties bevatten geavanceerde detailhandelsprijzen en promoties, catalogi, geschenkbonnen, loyaliteitsprogramma's en coupons.</span><span class="sxs-lookup"><span data-stu-id="4d78a-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="4d78a-107">Callcenterorders worden ook gebruikt door de POS-toepassing (Point of Sales) ter ondersteuning van afhandelingsscenario's van orders tussen afzetkanalen.</span><span class="sxs-lookup"><span data-stu-id="4d78a-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="4d78a-108">Het is belangrijk te weten dat de callcentermodule kan worden gebruikt door andere bedrijfstakken dan de detailhandel, maar de huidige versie van de toepassing Dynamics 365 voor Retail-callcenter is niet geoptimaliseerd voor gebruik in B2B-orderverwerkingsscenario´s of scenario's waarin orders een grote hoeveelheid verkoopregels hebben.</span><span class="sxs-lookup"><span data-stu-id="4d78a-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Dynamics 365 for Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="4d78a-109">Het is raadzaam dat gebruikers die gebruik willen maken van de callcenterfuncties voor orderverwerking buiten de verwerking van rechtstreekse transacties met de consument, voldoende tijd nemen om te testen en te valideren of activering van de callcenterfunctionaliteit voldoet aan functionele en prestatievereisten.</span><span class="sxs-lookup"><span data-stu-id="4d78a-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="4d78a-110">Met de callcentermodule kunnen orders worden gemaakt en wordt een gebruiksvriendelijke klantservicetoepassing geleverd die het eenvoudiger maakt voor gebruikers om klantaccounts te vinden en om alle gerelateerde klantordergegevens en -kenmerken te controleren.</span><span class="sxs-lookup"><span data-stu-id="4d78a-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="4d78a-111">Het klantservicescherm is ontworpen om een gebruiker snel toegang te verschaffen tot ordergerelateerde gegevens waarmee de meest voorkomende ordergerelateerde vragen worden beantwoord die van klanten worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="4d78a-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="4d78a-112">Deze pagina bevat koppelingen naar relevante documentatie met betrekking tot de installatie, configuratie en het functionele gebruik van de callcenterfuncties in Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="4d78a-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Dynamics 365 for Retail.</span></span>

## <a name="configure-the-call-center"></a><span data-ttu-id="4d78a-113">Het callcenter configureren</span><span class="sxs-lookup"><span data-stu-id="4d78a-113">Configure the call center</span></span>
[<span data-ttu-id="4d78a-114">Orderverwerkingsopties instellen</span><span class="sxs-lookup"><span data-stu-id="4d78a-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="4d78a-115">Orderverwerking configureren</span><span class="sxs-lookup"><span data-stu-id="4d78a-115">Configure order processing</span></span>
[<span data-ttu-id="4d78a-116">Fraudewaarschuwingen instellen</span><span class="sxs-lookup"><span data-stu-id="4d78a-116">Set up fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="4d78a-117">Handmatige orderwachtstanden</span><span class="sxs-lookup"><span data-stu-id="4d78a-117">Manual Order Holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="4d78a-118">Betalingsverwerking configureren</span><span class="sxs-lookup"><span data-stu-id="4d78a-118">Configure payment processing</span></span>
[<span data-ttu-id="4d78a-119">Betalingsmethoden in een callcenter</span><span class="sxs-lookup"><span data-stu-id="4d78a-119">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="4d78a-120">Leveringsmethoden configureren</span><span class="sxs-lookup"><span data-stu-id="4d78a-120">Configure delivery modes</span></span>
[<span data-ttu-id="4d78a-121">Leveringsmethoden en toeslagen van callcenters configureren</span><span class="sxs-lookup"><span data-stu-id="4d78a-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="4d78a-122">Direct marketing configureren</span><span class="sxs-lookup"><span data-stu-id="4d78a-122">Configure direct marketing</span></span>
[<span data-ttu-id="4d78a-123">Callcentercatalogi</span><span class="sxs-lookup"><span data-stu-id="4d78a-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="4d78a-124">RFM-analyse instellen</span><span class="sxs-lookup"><span data-stu-id="4d78a-124">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="4d78a-125">Continuïteitsprogramma's configureren</span><span class="sxs-lookup"><span data-stu-id="4d78a-125">Configure continuity programs</span></span>
[<span data-ttu-id="4d78a-126">Een continuïteitsprogramma instellen voor een callcenter</span><span class="sxs-lookup"><span data-stu-id="4d78a-126">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)


