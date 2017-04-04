---
title: Inkooporders voor een project
description: Dit artikel beschrijft de verschillende methoden die u kunt gebruiken om inkooporders voor een project te maken. De methode die u gebruikt, wordt bepaald door het doel van de inkooporder, wanneer de gekochte artikelen worden verbruikt, en wanneer ze bij een project in rekening worden gebracht.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 82305cfe38e7193cece3b9e7784fb81fd40f9c70
ms.lasthandoff: 03/31/2017


---

# <a name="purchase-orders-for-a-project"></a>Inkooporders voor een project

Dit artikel beschrijft de verschillende methoden die u kunt gebruiken om inkooporders voor een project te maken. De methode die u gebruikt, wordt bepaald door het doel van de inkooporder, wanneer de gekochte artikelen worden verbruikt, en wanneer ze bij een project in rekening worden gebracht.

In Microsoft Dynamics 365 voor bewerkingen, kunt u meerdere methoden gebruiken om inkooporders voor een project te maken. De methode die u gebruikt, wordt bepaald door het doel van de inkooporder, wanneer de gekochte artikelen worden verbruikt, en wanneer ze bij een project in rekening worden gebracht.

### <a name="methods-for-creating-a-purchase-order"></a>Methoden voor de aanmaak van een inkooporder

U kunt op een van de volgende manieren een inkooporder in Projectbeheer en boekhouding maken. Het doel van de inkooporder bepaalt wanneer de inkooporder wordt verbruikt en dus wanneer artikelen bij een project in rekening worden gebracht.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Methode</th>
<th>Doel</th>
<th>Verbruik van artikelen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Een inkooporder maken, direct van een project</td>
<td>Gebruik deze methode om artikelen van een externe leverancier voor verbruik bij een project te kopen. U kunt de inkooporder op twee manieren maken:
<ul>
<li>Vanuit het project zelf. In dit geval is het project al voor de inkooporder gedefinieerd.</li>
<li>Door naar de projectinkooporder te navigeren. U moet zowel de leverancier als het project selecteren waarvoor de inkooporder moet worden gemaakt.</li>
</ul></td>
<td>Artikelen die worden verbruikt wanneer de leveranciersfactuur wordt bijgewerkt.</td>
</tr>
<tr class="even">
<td>Een inkooporder van een verkooporder maken.</td>
<td>Gebruik deze methode om artikelen te kopen wanneer u een verkooporder van een project maakt.</td>
<td>Artikelen worden verbruikt wanneer de verkooporder bij de klant wordt gefactureerd.</td>
</tr>
<tr class="odd">
<td>Een inkooporder van een artikelbehoefte maken.</td>
<td>Gebruik deze methode om artikelen te kopen wanneer u een artikelbehoefte van een project maakt.</td>
<td>Artikelen worden verbruikt wanneer de pakbon van de artikelbehoefte wordt bijgewerkt.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Wanneer u de leveranciersfactuur of pakbon bijwerkt, wordt u gevraagd de pakbon op de artikelbehoefte te werken.


