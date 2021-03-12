---
title: Overzicht van Transportbeheer
description: Dit onderwerp bevat een overzicht van de functionaliteit voor transportbeheer in Supply Chain Management.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench, TMSLoadBuildTemplateApply, WHSLoadTemplate, TMSTransportationStatus, TMSLoadSeal, TMSLoadBuildProposal, TMSLoadBuildWorkbench, TMSLoadBuildStrategy, TMSLoadBuildStrategyAttributeValue
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fca83ef2c80ed6df9cfbdedd2805e453df3f737a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006486"
---
# <a name="transportation-management-overview"></a>Overzicht van Transportbeheer

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat een overzicht van de functionaliteit voor transportbeheer in Supply Chain Management.

Met Transportbeheer kunt u het transport van uw bedrijf gebruiken en kunt u tevens leveranciers- en routeringoplossingen voor binnenkomende en uitgaande orders identificeren. Bijvoorbeeld, kunt u de snelste route of het minste dure tarief voor een zending identificeren. In de volgende tabel worden de hoofdscenario´s beschreven voor het gebruik van Transportbeheer.

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
<td>Het eigen wagenpark van het bedrijf is beschikbaar voor levering/ophalen en de leveringstoeslagen worden doorberekend aan de klanten.</td>
<td>Voor de uitgaande processen kunt u Transportbeheer gebruiken om de transporttoeslagen te bepalen en deze door te berekenen aan klanten. Het factuurafstemmingsproces van de vervoerder is echter niet vereist.</td>
</tr>
<tr class="odd">
<td>Het eigen wagenpark van het bedrijf is beschikbaar voor levering/ophalen, maar de leveringstoeslagen worden niet doorberekend aan klanten, omdat de productprijzen inclusief transport zijn.</td>
<td>Veel van de functionaliteit Transportbeheer is niet vereist. U kunt Transportbeheer echter gebruiken om de transporttarieven te bepalen en de verkoopprijs dienovereenkomstig aan te passen.</td>
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

## <a name="planning-transportation-in-supply-chain-management"></a>Transport plannen in Supply Chain Management
In Transportbeheer kan transportplanning worden gebaseerd op orders of op verzendingen die zijn gemaakt op basis van deze orders. De verzendingen vinden altijd op een bepaald punt in de tijd plaats, maar zijn niet voor transportplanning vereist. De transferorders maken deel uit van het uitgaande scenario en kunnen samen met verkooporders worden gepland. 

![Ladingtekening](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Binnenkomend transport
Wanneer u artikelen bestelt bij een leverancier en deze in uw magazijn moeten worden geleverd, kunt u bijvoorbeeld het transport van de artikelen zelf bepalen. U kunt Supply Chain Management gebruiken om het transport en de ontvangst van een inkomende lading te plannen. De volgende afbeelding toont het bedrijfs processtroom voor het plannen van een verzending voor een binnenkomende lading. 

![Bedrijfsprocesstroom voor binnenkomend ladingtransport](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Uitgaand transport
U kunt een uitgaande lading plannen en verwerken om specifieke artikelen te verzenden van het magazijn van een bedrijf naar een klant. U kunt Supply Chain Management gebruiken om het transport en de verzending van een uitgaande lading te plannen. De volgende afbeelding toont de bedrijfsprocesstroom voor het plannen en verwerken van uitgaande lading voor verzending. 

![Uitgaande ladingen plannen en verwerken](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Lading opbouwen
Supply Chain Management bevat een strategie voor het opbouwen van ladingen die de op volume gebaseerde ladingopbouwstrategie wordt genoemd. Met deze strategie kunt u de maximumwaarden gebruiken die worden opgegeven voor hoogte en gewicht in de ladingsjabloon. U kunt ook de instellingen overschrijven door nieuwe waarden in te voeren. Als u deze strategie wilt gebruiken, selecteert u deze in het veld **Ladingopbouwstrategie** op het sneltabblad **Instellen** in het formulier **Workbench voor ladingopbouw**. Bovendien kunt u uw eigen belasting-bouwende strategieën toevoegen door een nieuwe klasse in de Application Object Tree (AOT) te maken.



