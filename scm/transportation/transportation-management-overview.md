---
title: Overzicht van Transportbeheer
description: Dit onderwerp bevat een overzicht van de functionaliteit voor het transport in Microsoft Dynamics 365 for Operations.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3136fd95c4c56495a391668d6c854a6ae1e36479
ms.lasthandoff: 03/31/2017


---

# <a name="transportation-management-overview"></a>Overzicht van Transportbeheer

Dit onderwerp bevat een overzicht van de functionaliteit voor het transport in Microsoft Dynamics 365 for Operations.

Met Transportbeheer kunt u het transport van uw bedrijf beheren en kunt u tevens leveranciers- en routeringoplossingen voor binnenkomende en uitgaande orders identificeren. Bijvoorbeeld, kunt u de snelste route of het minste dure tarief voor een zending identificeren. In de volgende tabel worden de hoofdscenario´s beschreven voor het gebruik van Transportbeheer in Microsoft Dynamics 365 for Operations.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenario</th>
<th>Gebruik van transportbeheer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Providers van externe logistiek voor transportactiviteiten gebruiken.</td>
<td>Transportbeheer voor binnenkomend en uitgaand transport gebruiken.</td>
</tr>
<tr class="even">
<td>Het eigen wagenpark van het bedrijf is beschikbaar voor levering/ophalen en de leveringstoeslagen worden doorberekend aan de klanten.</td>
<td>Voor de uitgaande processen kunt u Transportbeheer gebruiken om de transporttoeslagen te bepalen en deze door te berekenen aan klanten. Het factuurafstemmingsproces van de vervoerder is echter niet vereist.</td>
</tr>
<tr class="odd">
<td>Het eigen wagenpark van het bedrijf is beschikbaar voor levering/ophalen, maar de leveringstoeslagen worden niet doorberekend aan klanten, omdat de productprijzen inclusief transport zijn.</td>
<td>Veel van de functionaliteit Transportbeheer is niet vereist. U kunt Transportbeheer echter gebruiken om de transporttarieven te bepalen en de verkoopprijs dienovereenkomstig aan te passen.</td>
</tr>
<tr class="even">
<td>De logistieke service wordt door een andere rechtspersoon in hetzelfde bedrijf verleend.</td>
<td><ul>
<li>U kunt Transportbeheer gebruiken door de andere rechtspersoon als een andere vervoerder te behandelen. U kunt de economische transacties tussen rechtspersonen niet automatiseren. Daarom moet u deze handmatig transacties handmatig verwerken (bijvoorbeeld door een inkooporder te maken).</li>
<li>In de rechtspersoon die de logistieke services aanbiedt kan Transportbeheer worden gebruikt om transporttarieven te bepalen.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-dynamics-365-for-operations"></a>Planningstransport in Dynamics 365 for Operations
In Transportbeheer kan transportplanning worden gebaseerd op orders of op verzendingen die zijn gemaakt op basis van deze orders. De verzendingen vinden altijd op een bepaald punt in de tijd plaats, maar zijn niet voor transportplanning vereist. De transferorders maken deel uit van het uitgaande scenario en kunnen samen met verkooporders worden gepland. 

![Tekening laden](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Binnenkomend transport
Wanneer u artikelen bij een leverancier bestelt en de artikelen moeten worden geleverd op uw magazijn, is het raadzaam om te bepalen of het transport van de artikelen zelf. Dynamics 365 for Operations kunt u van plan bent de transport- en ontvangst van de inkomende belasting. De volgende afbeelding toont het bedrijfs processtroom voor het plannen van een verzending voor een binnenkomende lading. 

![Bedrijfsprocesstroom voor binnenkomend ladingtransport](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Uitgaand transport
U kunt een uitgaande lading plannen en verwerken om specifieke artikelen te verzenden van het magazijn van een bedrijf naar een klant. U kunt Dynamics 365 for Operations gebruiken om het transport en de verzending van een uitgaande lading te plannen. De volgende afbeelding toont de bedrijfsprocesstroom voor het plannen en verwerken van uitgaande lading voor verzending. 

![Planning en het verwerken van uitgaande wordt geladen](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Lading opbouwen
Dynamics 365 for Operations bevat een strategie voor het opbouwen van ladingen die de op volume gebaseerde ladingopbouwstrategie wordt genoemd. Met deze strategie kunt u de maximumwaarden gebruiken die worden opgegeven voor hoogte en gewicht in de ladingsjabloon. U kunt ook de instellingen overschrijven door nieuwe waarden in te voeren. Als u deze strategie wilt gebruiken, selecteert u deze in het veld **Ladingopbouwstrategie** op het sneltabblad **Instellen** in het formulier **Workbench voor ladingopbouw**. Bovendien kunt u uw eigen belasting-bouwende strategieën toevoegen door een nieuwe klasse in de Application Object Tree (AOT) te maken.


