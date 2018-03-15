---
title: Inkooporders voor een project
description: Dit artikel beschrijft de verschillende methoden die u kunt gebruiken om inkooporders voor een project te maken. De methode die u gebruikt, wordt bepaald door het doel van de inkooporder, wanneer de gekochte artikelen worden verbruikt, en wanneer ze bij een project in rekening worden gebracht.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 1797bc49877f1c8c06797083d1c7b76934675ba3
ms.contentlocale: nl-nl
ms.lasthandoff: 02/07/2018

---

# <a name="purchase-orders-for-a-project"></a>Inkooporders voor een project

[!include[banner](../includes/banner.md)]


Dit artikel beschrijft de verschillende methoden die u kunt gebruiken om inkooporders voor een project te maken. De methode die u gebruikt, wordt bepaald door het doel van de inkooporder, wanneer de gekochte artikelen worden verbruikt, en wanneer ze bij een project in rekening worden gebracht.

In Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, kunt u meerdere methoden gebruiken om inkooporders voor een project te maken. De methode die u gebruikt, wordt bepaald door het doel van de inkooporder, wanneer de gekochte artikelen worden verbruikt, en wanneer ze bij een project in rekening worden gebracht.

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
> Wanneer u de leveranciersfactuur of pakbon bijwerkt, wordt u gevraagd de pakbon op de artikelbehoefte bij te werken.

Zie [Artikelen ontvangen op een inkooporder vanuit een artikelbehoefte](tasks/receive-items-purchase-order-item-requirement.md) voor meer informatie.


