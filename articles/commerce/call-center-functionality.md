---
title: Verkoopfunctionaliteit callcenter
description: Dit onderwerp bevat een overzicht van de functionaliteit voor callcenterverkoop in Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 816bfc8b93f52fe91192874bcc1c8e605e41b582
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022097"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="19948-103">Verkoopfunctionaliteit callcenter</span><span class="sxs-lookup"><span data-stu-id="19948-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="19948-104">In Dynamics 365 Commerce is een callcenter een type afzetkanaal dat kan worden gedefinieerd in de toepassing.</span><span class="sxs-lookup"><span data-stu-id="19948-104">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="19948-105">Als u een specifiek kanaal definieert voor uw callcenterentiteiten, kan het systeem specifieke gegevensstandaardwaarden en standaardwaarden voor orderverwerking koppelen aan verkooporders die zijn gemaakt door een gebruiker of het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="19948-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="19948-106">Callcenterfuncties bevatten geavanceerde prijzen en promoties, catalogi, geschenkbonnen, loyaliteitsprogramma's en coupons.</span><span class="sxs-lookup"><span data-stu-id="19948-106">Call center features include advanced price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="19948-107">Callcenterorders worden ook gebruikt door de POS-toepassing (Point of Sales) ter ondersteuning van afhandelingsscenario's van orders tussen afzetkanalen.</span><span class="sxs-lookup"><span data-stu-id="19948-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="19948-108">Het is belangrijk te weten dat de callcentermodule kan worden gebruikt door andere bedrijfstakken dan Commerce, maar de huidige versie van de toepassing -callcenter is niet geoptimaliseerd voor gebruik in B2B-orderverwerkingsscenario's of scenario's waarin orders een grote hoeveelheid verkoopregels hebben.</span><span class="sxs-lookup"><span data-stu-id="19948-108">It's important to note that while the call center module can be utilized by other industries outside of Commerce, the current release of the call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="19948-109">Het is raadzaam dat gebruikers die gebruik willen maken van de callcenterfuncties voor orderverwerking buiten de verwerking van rechtstreekse transacties met de consument, voldoende tijd nemen om te testen en te valideren of activering van de callcenterfunctionaliteit voldoet aan functionele en prestatievereisten.</span><span class="sxs-lookup"><span data-stu-id="19948-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="19948-110">Met de callcentermodule kunnen orders worden gemaakt en wordt een gebruiksvriendelijke klantservicetoepassing geleverd die het eenvoudiger maakt voor gebruikers om klantaccounts te vinden en om alle gerelateerde klantordergegevens en -kenmerken te controleren.</span><span class="sxs-lookup"><span data-stu-id="19948-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="19948-111">Het klantservicescherm is ontworpen om een gebruiker snel toegang te verschaffen tot ordergerelateerde gegevens waarmee de meest voorkomende ordergerelateerde vragen worden beantwoord die van klanten worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="19948-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="19948-112">Deze pagina bevat koppelingen naar relevante documentatie met betrekking tot de installatie, configuratie en het functionele gebruik van de callcenterfuncties.</span><span class="sxs-lookup"><span data-stu-id="19948-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="19948-113">Het callcenter configureren</span><span class="sxs-lookup"><span data-stu-id="19948-113">Configure the call center</span></span>

[<span data-ttu-id="19948-114">Callcenterkanalen instellen</span><span class="sxs-lookup"><span data-stu-id="19948-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="19948-115">Orderverwerking configureren</span><span class="sxs-lookup"><span data-stu-id="19948-115">Configure order processing</span></span>

[<span data-ttu-id="19948-116">Fraudewaarschuwingen van callcenters instellen en gebruiken</span><span class="sxs-lookup"><span data-stu-id="19948-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="19948-117">Configureren en werken met orderwachtstanden voor callcenters</span><span class="sxs-lookup"><span data-stu-id="19948-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="19948-118">Betalingsverwerking configureren</span><span class="sxs-lookup"><span data-stu-id="19948-118">Configure payment processing</span></span>

[<span data-ttu-id="19948-119">Betalingsmethoden in callcenters</span><span class="sxs-lookup"><span data-stu-id="19948-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="19948-120">Leveringsmethoden configureren</span><span class="sxs-lookup"><span data-stu-id="19948-120">Configure delivery modes</span></span>

[<span data-ttu-id="19948-121">Leveringsmethoden en toeslagen van callcenters configureren</span><span class="sxs-lookup"><span data-stu-id="19948-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="19948-122">Direct marketing configureren</span><span class="sxs-lookup"><span data-stu-id="19948-122">Configure direct marketing</span></span>

[<span data-ttu-id="19948-123">Callcentercatalogi</span><span class="sxs-lookup"><span data-stu-id="19948-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="19948-124">Recency-, frequentie- en monetaire analyse (RFM) instellen</span><span class="sxs-lookup"><span data-stu-id="19948-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="19948-125">Continuïteitsprogramma's configureren</span><span class="sxs-lookup"><span data-stu-id="19948-125">Configure continuity programs</span></span>

[<span data-ttu-id="19948-126">Continuïteitsprogramma's instellen voor callcenters</span><span class="sxs-lookup"><span data-stu-id="19948-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
