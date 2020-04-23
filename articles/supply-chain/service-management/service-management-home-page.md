---
title: Overzicht van Servicebeheer
description: Met Servicebeheer kunt u serviceovereenkomsten en serviceabonnementen vastleggen, serviceorders en vragen van klanten afhandelen en de levering van services aan klanten beheren en analyseren.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c58cd8002f6bb80ebcbd8c552e4e3509d7528ea
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215166"
---
# <a name="service-management-overview"></a><span data-ttu-id="456d4-103">Overzicht van Servicebeheer</span><span class="sxs-lookup"><span data-stu-id="456d4-103">Service management overview</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="456d4-104">Met **Servicebeheer** kunt u serviceovereenkomsten en serviceabonnementen vastleggen, serviceorders en vragen van klanten afhandelen en de levering van services aan klanten beheren en analyseren.</span><span class="sxs-lookup"><span data-stu-id="456d4-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="456d4-105">Met serviceovereenkomsten kunt u de resources opgeven die bij een standaardonderhoudsbezoek worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="456d4-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="456d4-106">Daarnaast kunt u serviceovereenkomsten gebruiken om te bekijken hoe deze resources worden gefactureerd aan de klant.</span><span class="sxs-lookup"><span data-stu-id="456d4-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="456d4-107">Een serviceovereenkomst kan ook een serviceovereenkomst bevatten waarmee standaardreactietijden worden opgegeven en die functies bevat voor het vastleggen van de werkelijke tijd.</span><span class="sxs-lookup"><span data-stu-id="456d4-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="456d4-108">U kunt serviceorders maken om informatie over geplande en ongeplande bezoeken door een onderhoudsmonteur aan een klant te beheren.</span><span class="sxs-lookup"><span data-stu-id="456d4-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="456d4-109">Serviceorders bevatten onder andere de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="456d4-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="456d4-110">Het aantal uren werk dat de onderhoudsmonteur uitvoert</span><span class="sxs-lookup"><span data-stu-id="456d4-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="456d4-111">Het type onderhoud of reparatie</span><span class="sxs-lookup"><span data-stu-id="456d4-111">The type of service or repair</span></span>

3.  <span data-ttu-id="456d4-112">Het artikel dat moet worden gerepareerd, inclusief details over de symptomen en de diagnose</span><span class="sxs-lookup"><span data-stu-id="456d4-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="456d4-113">Onkosten en bijzondere kosten die zijn gerelateerd aan het onderhoud of de reparatie</span><span class="sxs-lookup"><span data-stu-id="456d4-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="456d4-114">U kunt serviceaanvragen ontvangen, verwerken en verzenden.</span><span class="sxs-lookup"><span data-stu-id="456d4-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="456d4-115">Wanneer u een serviceorder hebt gemaakt, kunt u servicefasen gebruiken om de voortgang te controleren en kunt u regels opgeven waarmee wordt bepaald welke acties zijn ingeschakeld in elke fase.</span><span class="sxs-lookup"><span data-stu-id="456d4-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="456d4-116">Wanneer een serviceorder is voltooid, kunt u afmelden op de order om te bevestigen dat deze is voltooid. Vervolgens kunt u de order boeken om het factureringsproces te starten.</span><span class="sxs-lookup"><span data-stu-id="456d4-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="456d4-117">Met de rapportagefunctie kunt u serviceordermarges en abonnementstransacties controleren en werkomschrijvingen en -ontvangsten afdrukken.</span><span class="sxs-lookup"><span data-stu-id="456d4-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="456d4-118">Bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="456d4-118">Business processes</span></span>

<span data-ttu-id="456d4-119">In het volgende diagram worden de bedrijfsprocessen op hoog niveau voor **Servicebeheer** aangegeven en wordt weergegeven waar de serviceprocessen zijn geïntegreerd met andere modules.</span><span class="sxs-lookup"><span data-stu-id="456d4-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules.</span></span>

<span data-ttu-id="456d4-120">[![Diagram van bedrijfsproces Servicebeheer](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="456d4-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="456d4-121">Servicebeheer in één oogopslag</span><span class="sxs-lookup"><span data-stu-id="456d4-121">Service management at a glance</span></span>

|<span data-ttu-id="456d4-122">Belangrijke taken</span><span class="sxs-lookup"><span data-stu-id="456d4-122">Important tasks</span></span>           | <span data-ttu-id="456d4-123">Primaire pagina's</span><span class="sxs-lookup"><span data-stu-id="456d4-123">Primary pages</span></span>                         |<span data-ttu-id="456d4-124">Veelgebruikte rapporten</span><span class="sxs-lookup"><span data-stu-id="456d4-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="456d4-125">Serviceovereenkomsten uitvoeren</span><span class="sxs-lookup"><span data-stu-id="456d4-125">Fulfill service agreements</span></span>|<span data-ttu-id="456d4-126">Serviceovereenkomsten</span><span class="sxs-lookup"><span data-stu-id="456d4-126">Service agreements</span></span>                     |<span data-ttu-id="456d4-127">Marge van serviceorder</span><span class="sxs-lookup"><span data-stu-id="456d4-127">Service order margin</span></span>         |
|<span data-ttu-id="456d4-128">Vragen van klanten afhandelen</span><span class="sxs-lookup"><span data-stu-id="456d4-128">Handle customer inquiries</span></span> |<span data-ttu-id="456d4-129">Serviceorders</span><span class="sxs-lookup"><span data-stu-id="456d4-129">Service orders</span></span>                         |<span data-ttu-id="456d4-130">Werkomschrijving</span><span class="sxs-lookup"><span data-stu-id="456d4-130">Work description</span></span>             |
|                          |<span data-ttu-id="456d4-131">Verzendbord</span><span class="sxs-lookup"><span data-stu-id="456d4-131">Dispatch board</span></span>                         |<span data-ttu-id="456d4-132">Transactie - abonnement</span><span class="sxs-lookup"><span data-stu-id="456d4-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="456d4-133">Abonnementskostentransacties</span><span class="sxs-lookup"><span data-stu-id="456d4-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="456d4-134">Integratie van Servicebeheer</span><span class="sxs-lookup"><span data-stu-id="456d4-134">Integration of Service management</span></span>

<span data-ttu-id="456d4-135">Servicebeheer kan worden geïntegreerd met de volgende modules:</span><span class="sxs-lookup"><span data-stu-id="456d4-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="456d4-136">Overzicht van Verkoop en marketing</span><span class="sxs-lookup"><span data-stu-id="456d4-136">Sales and marketing overview</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="456d4-137">Human Resources</span><span class="sxs-lookup"><span data-stu-id="456d4-137">Human resources</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/index)

  

