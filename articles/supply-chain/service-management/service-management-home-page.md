---
title: Servicebeheer
description: Met Servicebeheer kunt u serviceovereenkomsten en serviceabonnementen vastleggen, serviceorders en vragen van klanten afhandelen en de levering van services aan klanten beheren en analyseren.
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: nl-nl
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="80a69-103">Servicebeheer</span><span class="sxs-lookup"><span data-stu-id="80a69-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="80a69-104">Met **Servicebeheer** kunt u serviceovereenkomsten en serviceabonnementen vastleggen, serviceorders en vragen van klanten afhandelen en de levering van services aan klanten beheren en analyseren.</span><span class="sxs-lookup"><span data-stu-id="80a69-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="80a69-105">Met serviceovereenkomsten kunt u de resources opgeven die bij een standaardonderhoudsbezoek worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="80a69-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="80a69-106">Daarnaast kunt u serviceovereenkomsten gebruiken om te bekijken hoe deze resources worden gefactureerd aan de klant.</span><span class="sxs-lookup"><span data-stu-id="80a69-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="80a69-107">Een serviceovereenkomst kan ook een serviceovereenkomst bevatten waarmee standaardreactietijden worden opgegeven en die functies bevat voor het vastleggen van de werkelijke tijd.</span><span class="sxs-lookup"><span data-stu-id="80a69-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="80a69-108">U kunt serviceorders maken om informatie over geplande en ongeplande bezoeken door een onderhoudsmonteur aan een klant te beheren.</span><span class="sxs-lookup"><span data-stu-id="80a69-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="80a69-109">Serviceorders bevatten onder andere de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="80a69-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="80a69-110">Het aantal uren werk dat de onderhoudsmonteur uitvoert</span><span class="sxs-lookup"><span data-stu-id="80a69-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="80a69-111">Het type onderhoud of reparatie</span><span class="sxs-lookup"><span data-stu-id="80a69-111">The type of service or repair</span></span>

3.  <span data-ttu-id="80a69-112">Het artikel dat moet worden gerepareerd, inclusief details over de symptomen en de diagnose</span><span class="sxs-lookup"><span data-stu-id="80a69-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="80a69-113">Onkosten en bijzondere kosten die zijn gerelateerd aan het onderhoud of de reparatie</span><span class="sxs-lookup"><span data-stu-id="80a69-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="80a69-114">Klanten kunnen serviceaanvragen indienen via internet met de Enterprise Portal.</span><span class="sxs-lookup"><span data-stu-id="80a69-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="80a69-115">U kunt deze aanvragen ontvangen, verwerken en verzenden.</span><span class="sxs-lookup"><span data-stu-id="80a69-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="80a69-116">Wanneer u een serviceorder hebt gemaakt, kunt u servicefasen gebruiken om de voortgang te controleren en kunt u regels opgeven waarmee wordt bepaald welke acties zijn ingeschakeld in elke fase.</span><span class="sxs-lookup"><span data-stu-id="80a69-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="80a69-117">Wanneer een serviceorder is voltooid, kunt u afmelden op de order om te bevestigen dat deze is voltooid. Vervolgens kunt u de order boeken om het factureringsproces te starten.</span><span class="sxs-lookup"><span data-stu-id="80a69-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="80a69-118">Met de rapportagefunctie kunt u serviceordermarges en abonnementstransacties controleren en werkomschrijvingen en -ontvangsten afdrukken.</span><span class="sxs-lookup"><span data-stu-id="80a69-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="80a69-119">Bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="80a69-119">Business processes</span></span>

<span data-ttu-id="80a69-120">In het volgende diagram worden de bedrijfsprocessen op hoog niveau voor **Servicebeheer** aangegeven en wordt weergegeven waar de serviceprocessen zijn geïntegreerd met andere modules in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="80a69-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="80a69-121">[![Diagram van bedrijfsproces Servicebeheer](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="80a69-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="80a69-122">Servicebeheer in één oogopslag</span><span class="sxs-lookup"><span data-stu-id="80a69-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80a69-123">Belangrijke taken</span><span class="sxs-lookup"><span data-stu-id="80a69-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="80a69-124">Primaire formulieren</span><span class="sxs-lookup"><span data-stu-id="80a69-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="80a69-125">Veelgebruikte rapporten</span><span class="sxs-lookup"><span data-stu-id="80a69-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80a69-126">Serviceovereenkomsten uitvoeren</span><span class="sxs-lookup"><span data-stu-id="80a69-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="80a69-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Serviceovereenkomsten (formulier)</a></span><span class="sxs-lookup"><span data-stu-id="80a69-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="80a69-128"><strong>Marge van serviceorder</strong></span><span class="sxs-lookup"><span data-stu-id="80a69-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80a69-129">Vragen van klanten afhandelen</span><span class="sxs-lookup"><span data-stu-id="80a69-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="80a69-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Serviceorders (formulier)</a></span><span class="sxs-lookup"><span data-stu-id="80a69-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="80a69-131"><strong>Werkomschrijving</strong></span><span class="sxs-lookup"><span data-stu-id="80a69-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="80a69-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Verzendbord (formulier)</a></span><span class="sxs-lookup"><span data-stu-id="80a69-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="80a69-133"><strong>Transactie - abonnement</strong></span><span class="sxs-lookup"><span data-stu-id="80a69-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="80a69-134"><strong>Abonnementskostentransacties</strong></span><span class="sxs-lookup"><span data-stu-id="80a69-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="80a69-135">Integratie van Servicebeheer</span><span class="sxs-lookup"><span data-stu-id="80a69-135">Integration of Service management</span></span>

<span data-ttu-id="80a69-136">Servicebeheer kan worden geïntegreerd met de volgende modules in Microsoft Dynamics 365 for Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="80a69-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="80a69-137">Verkoop en marketing</span><span class="sxs-lookup"><span data-stu-id="80a69-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="80a69-138">HRM</span><span class="sxs-lookup"><span data-stu-id="80a69-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


