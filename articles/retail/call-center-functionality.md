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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e85b65e116b32adca09e46252d7d3bbe5101e1cf
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="call-center"></a><span data-ttu-id="e8dbb-103">Callcenter</span><span class="sxs-lookup"><span data-stu-id="e8dbb-103">Call center</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="e8dbb-104">In Dynamics 365 for Retail is een callcenter een type detailhandelafzetkanaal dat kan worden gedefinieerd in de toepassing.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-104">In Dynamics 365 for Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="e8dbb-105">Als u een specifiek kanaal definieert voor uw callcenterentiteiten, kan het systeem specifieke gegevensstandaardwaarden en standaardwaarden voor orderverwerking koppelen aan verkooporders die zijn gemaakt door een gebruiker of het callcenterkanaal.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="e8dbb-106">Callcenterfuncties bevatten geavanceerde detailhandelsprijzen en promoties, catalogi, geschenkbonnen, loyaliteitsprogramma's en coupons.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="e8dbb-107">Callcenterorders worden ook gebruikt door de POS-toepassing (Point of Sales) ter ondersteuning van afhandelingsscenario's van orders tussen afzetkanalen.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="e8dbb-108">Het is belangrijk te weten dat de callcentermodule kan worden gebruikt door andere bedrijfstakken dan de detailhandel, maar de huidige versie van de toepassing Dynamics 365 voor Retail-callcenter is niet geoptimaliseerd voor gebruik in B2B-orderverwerkingsscenario´s of scenario's waarin orders een grote hoeveelheid verkoopregels hebben.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Dynamics 365 for Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="e8dbb-109">Het is raadzaam dat gebruikers die gebruik willen maken van de callcenterfuncties voor orderverwerking buiten de verwerking van rechtstreekse transacties met de consument, voldoende tijd nemen om te testen en te valideren of activering van de callcenterfunctionaliteit voldoet aan functionele en prestatievereisten.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="e8dbb-110">Met de callcentermodule kunnen orders worden gemaakt en wordt een gebruiksvriendelijke klantservicetoepassing geleverd die het eenvoudiger maakt voor gebruikers om klantaccounts te vinden en om alle gerelateerde klantordergegevens en -kenmerken te controleren.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="e8dbb-111">Het klantservicescherm is ontworpen om een gebruiker snel toegang te verschaffen tot ordergerelateerde gegevens waarmee de meest voorkomende ordergerelateerde vragen worden beantwoord die van klanten worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="e8dbb-112">Deze pagina bevat koppelingen naar relevante documentatie met betrekking tot de installatie, configuratie en het functionele gebruik van de callcenterfuncties in Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="e8dbb-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Dynamics 365 for Retail.</span></span>

## <a name="configure-the-call-center"></a><span data-ttu-id="e8dbb-113">Het callcenter configureren</span><span class="sxs-lookup"><span data-stu-id="e8dbb-113">Configure the call center</span></span>
[<span data-ttu-id="e8dbb-114">Orderverwerkingsopties instellen</span><span class="sxs-lookup"><span data-stu-id="e8dbb-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="e8dbb-115">Orderverwerking configureren</span><span class="sxs-lookup"><span data-stu-id="e8dbb-115">Configure order processing</span></span>
<span data-ttu-id="e8dbb-116">[Fraudewaarschuwingen instellen](set-up-fraud-alerts.md)
[Handmatige orderwachtstanden](work-with-order-holds.md)</span><span class="sxs-lookup"><span data-stu-id="e8dbb-116">[Set up fraud alerts](set-up-fraud-alerts.md)
[Manual Order Holds](work-with-order-holds.md)</span></span>

## <a name="configure-payment-processing"></a><span data-ttu-id="e8dbb-117">Betalingsverwerking configureren</span><span class="sxs-lookup"><span data-stu-id="e8dbb-117">Configure payment processing</span></span>
[<span data-ttu-id="e8dbb-118">Betalingsmethoden in een callcenter</span><span class="sxs-lookup"><span data-stu-id="e8dbb-118">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="e8dbb-119">Direct marketing configureren</span><span class="sxs-lookup"><span data-stu-id="e8dbb-119">Configure direct marketing</span></span>
[<span data-ttu-id="e8dbb-120">Callcentercatalogi</span><span class="sxs-lookup"><span data-stu-id="e8dbb-120">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="e8dbb-121">RFM-analyse instellen</span><span class="sxs-lookup"><span data-stu-id="e8dbb-121">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="e8dbb-122">Continuïteitsprogramma's configureren</span><span class="sxs-lookup"><span data-stu-id="e8dbb-122">Configure continuity programs</span></span>
[<span data-ttu-id="e8dbb-123">Een continuïteitsprogramma instellen voor een callcenter</span><span class="sxs-lookup"><span data-stu-id="e8dbb-123">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)


