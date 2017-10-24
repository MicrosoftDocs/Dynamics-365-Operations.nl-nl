---
title: Overzicht van Transportbeheer
description: Dit onderwerp bevat een overzicht van de functionaliteit voor het transport in Microsoft Dynamics 365 for Finance and Operations.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1c71c8f6c4f94342ac18cbfb7dfbc02ddb3f9f35
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="transportation-management-overview"></a><span data-ttu-id="114e0-103">Overzicht van Transportbeheer</span><span class="sxs-lookup"><span data-stu-id="114e0-103">Transportation management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="114e0-104">Dit onderwerp bevat een overzicht van de functionaliteit voor het transport in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="114e0-104">This topic gives an overview of the transportation management functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="114e0-105">Met Transportbeheer kunt u het transport van uw bedrijf gebruiken en kunt u tevens leveranciers- en routeringoplossingen voor binnenkomende en uitgaande orders identificeren.</span><span class="sxs-lookup"><span data-stu-id="114e0-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="114e0-106">Bijvoorbeeld, kunt u de snelste route of het minste dure tarief voor een zending identificeren.</span><span class="sxs-lookup"><span data-stu-id="114e0-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="114e0-107">In de volgende tabel worden de hoofdscenario's beschreven voor het gebruik van Transportbeheer in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="114e0-107">The following table describes the main scenarios for using Transportation management in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="114e0-108">Scenario</span><span class="sxs-lookup"><span data-stu-id="114e0-108">Scenario</span></span></th>
<th><span data-ttu-id="114e0-109">Gebruik van transportbeheer</span><span class="sxs-lookup"><span data-stu-id="114e0-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="114e0-110">Providers van externe logistiek voor transportactiviteiten gebruiken.</span><span class="sxs-lookup"><span data-stu-id="114e0-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="114e0-111">Transportbeheer voor binnenkomend en uitgaand transport gebruiken.</span><span class="sxs-lookup"><span data-stu-id="114e0-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="114e0-112">Het eigen wagenpark van het bedrijf is beschikbaar voor levering/ophalen en de leveringstoeslagen worden doorberekend aan de klanten.</span><span class="sxs-lookup"><span data-stu-id="114e0-112">The company's own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="114e0-113">Voor de uitgaande processen kunt u Transportbeheer gebruiken om de transporttoeslagen te bepalen en deze door te berekenen aan klanten.</span><span class="sxs-lookup"><span data-stu-id="114e0-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="114e0-114">Het factuurafstemmingsproces van de vervoerder is echter niet vereist.</span><span class="sxs-lookup"><span data-stu-id="114e0-114">However, the carrier invoice reconciliation process isn't required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="114e0-115">Het eigen wagenpark van het bedrijf is beschikbaar voor levering/ophalen, maar de leveringstoeslagen worden niet doorberekend aan klanten, omdat de productprijzen inclusief transport zijn.</span><span class="sxs-lookup"><span data-stu-id="114e0-115">The company's own fleet is available for delivery/pickup, but delivery charges aren't passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="114e0-116">Veel van de functionaliteit Transportbeheer is niet vereist.</span><span class="sxs-lookup"><span data-stu-id="114e0-116">A lot of the Transportation management functionality isn't required.</span></span> <span data-ttu-id="114e0-117">U kunt Transportbeheer echter gebruiken om de transporttarieven te bepalen en de verkoopprijs dienovereenkomstig aan te passen.</span><span class="sxs-lookup"><span data-stu-id="114e0-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="114e0-118">De logistieke service wordt door een andere rechtspersoon in hetzelfde bedrijf verleend.</span><span class="sxs-lookup"><span data-stu-id="114e0-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="114e0-119">U kunt Transportbeheer gebruiken door de andere rechtspersoon als een andere vervoerder te behandelen.</span><span class="sxs-lookup"><span data-stu-id="114e0-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="114e0-120">U kunt de economische transacties tussen rechtspersonen niet automatiseren.</span><span class="sxs-lookup"><span data-stu-id="114e0-120">You can't automate the economic transactions between legal entities.</span></span> <span data-ttu-id="114e0-121">Daarom moet u deze handmatig transacties handmatig verwerken (bijvoorbeeld door een inkooporder te maken).</span><span class="sxs-lookup"><span data-stu-id="114e0-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="114e0-122">In de rechtspersoon die de logistieke services aanbiedt kan Transportbeheer worden gebruikt om transporttarieven te bepalen.</span><span class="sxs-lookup"><span data-stu-id="114e0-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a><span data-ttu-id="114e0-123">Transportplanning in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="114e0-123">Planning transportation in Finance and Operations</span></span>
<span data-ttu-id="114e0-124">In Transportbeheer kan transportplanning worden gebaseerd op orders of op verzendingen die zijn gemaakt op basis van deze orders.</span><span class="sxs-lookup"><span data-stu-id="114e0-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="114e0-125">De verzendingen vinden altijd op een bepaald punt in de tijd plaats, maar zijn niet voor transportplanning vereist.</span><span class="sxs-lookup"><span data-stu-id="114e0-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="114e0-126">De transferorders maken deel uit van het uitgaande scenario en kunnen samen met verkooporders worden gepland.</span><span class="sxs-lookup"><span data-stu-id="114e0-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![Ladingtekening](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="114e0-128">Binnenkomend transport</span><span class="sxs-lookup"><span data-stu-id="114e0-128">Inbound transportation</span></span>
<span data-ttu-id="114e0-129">Wanneer u artikelen bestelt bij een leverancier en deze in uw magazijn moeten worden geleverd, kunt u bijvoorbeeld het transport van de artikelen zelf bepalen.</span><span class="sxs-lookup"><span data-stu-id="114e0-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="114e0-130">U kunt Finance and Operations gebruiken om het transport en de ontvangst van een inkomende lading te plannen.</span><span class="sxs-lookup"><span data-stu-id="114e0-130">You can use Finance and Operations to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="114e0-131">De volgende afbeelding toont het bedrijfs processtroom voor het plannen van een verzending voor een binnenkomende lading.</span><span class="sxs-lookup"><span data-stu-id="114e0-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![Bedrijfsprocesstroom voor binnenkomend ladingtransport](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="114e0-133">Uitgaand transport</span><span class="sxs-lookup"><span data-stu-id="114e0-133">Outbound transportation</span></span>
<span data-ttu-id="114e0-134">U kunt een uitgaande lading plannen en verwerken om specifieke artikelen te verzenden van het magazijn van een bedrijf naar een klant.</span><span class="sxs-lookup"><span data-stu-id="114e0-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="114e0-135">U kunt Finance and Operations gebruiken om het transport en de verzending van een uitgaande lading te plannen.</span><span class="sxs-lookup"><span data-stu-id="114e0-135">You can use Finance and Operations to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="114e0-136">De volgende afbeelding toont de bedrijfsprocesstroom voor het plannen en verwerken van uitgaande lading voor verzending.</span><span class="sxs-lookup"><span data-stu-id="114e0-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![Uitgaande ladingen plannen en verwerken](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="114e0-138">Lading opbouwen</span><span class="sxs-lookup"><span data-stu-id="114e0-138">Load building</span></span>
<span data-ttu-id="114e0-139">Finance and Operations bevat een strategie voor het opbouwen van ladingen die de op volume gebaseerde ladingopbouwstrategie wordt genoemd.</span><span class="sxs-lookup"><span data-stu-id="114e0-139">Finance and Operations provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="114e0-140">Met deze strategie kunt u de maximumwaarden gebruiken die worden opgegeven voor hoogte en gewicht in de ladingsjabloon. U kunt ook de instellingen overschrijven door nieuwe waarden in te voeren.</span><span class="sxs-lookup"><span data-stu-id="114e0-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="114e0-141">Als u deze strategie wilt gebruiken, selecteert u deze in het veld **Ladingopbouwstrategie** op het sneltabblad **Instellen** in het formulier **Workbench voor ladingopbouw**.</span><span class="sxs-lookup"><span data-stu-id="114e0-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="114e0-142">Bovendien kunt u uw eigen belasting-bouwende strategieën toevoegen door een nieuwe klasse in de Application Object Tree (AOT) te maken.</span><span class="sxs-lookup"><span data-stu-id="114e0-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>




