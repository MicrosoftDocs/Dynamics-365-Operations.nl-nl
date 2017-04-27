---
title: Waarden van voorraadobjecten
description: Dit artikel biedt informatie over hoe de waarden van een voorraadobject worden berekend.
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>Waarden van voorraadobjecten

Dit artikel biedt informatie over hoe de waarden van een voorraadobject worden berekend. 

Met een nieuwe functionaliteit die **fysieke hoeveelheid **wordt genoemd, kunt u de waarden van een specifiek voorraadobject zien. Een kostobject geeft het entiteitsniveau weer waarin de voorraadboekhouding wordt uitgevoerd. Voor meer informatie over kostenobjecten, zie [Kostenobjecten](cost-object.md). Om de waarden van een specifiek voorraadobject te bekijken, klikt u op **Fysieke hoeveelheid** op de pagina **Kostenobject**. De waarde van een voorraadobject wordt als volgt berekend: Voorraadobject.Waarde = Kostenobject.Gemiddelde eenheidskosten × Voorraadobject.Hoeveelheid. In het volgende voorbeeld zie u hoe de waarden van een voorraadobject en kostenobject worden berekend. Twee productontvangstbongebeurtenissen worden geregistreerd op artikel A:

-   Productontvangstbon 1: Hoeveelheid = 100 stuks, Bedrag = $ 1.000,00, Locatie = 1, Magazijn =11, Batchnr. = B1
-   Productontvangstbon 2: Hoeveelheid = 50 stuks, Bedrag = $ 800,00, Locatie = 1, Magazijn =11, Batchnr. = B2

De volgende tabel geeft het resultaat van de berekening voor een kostenobject. U kunt het resultaat op de pagina **Kostenobject** weergeven.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Objecttype</th>
<th>Artikelnummer</th>
<th>Locatie</th>
<th>Hoeveelheid</th>
<th>Voorraadeenheid</th>
<th>Waarde</th>
<th>Gemiddelde eenheidskosten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kostenobject</td>
<td>A</td>
<td>1</td>
<td>150</td>
<td>Stuks</td>
<td><p>$°1800,00</p></td>
<td><p>$°12,00</p></td>
</tr>
</tbody>
</table>

De volgende tabel geeft het resultaat van de berekening voor een voorraadobject. U kunt het resultaat bekijken door te klikken op **Fysieke hoeveelheid** op de pagina **Kostenobject**.

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Objecttype</th>
<th>Artikelnummer</th>
<th>Locatie</th>
<th>Magazijn</th>
<th>Batchnr.</th>
<th>Hoeveelheid</th>
<th>Voorraadeenheid</th>
<th>Waarde</th>
<th>Gemiddelde eenheidskosten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Voorraadobject</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>Stuks</td>
<td><p>$ 1200,00</p></td>
<td><p>$°12,00</p></td>
</tr>
<tr class="even">
<td>Voorraadobject</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>Stuks</td>
<td><p>$ 600,00</p></td>
<td><p>$°12,00</p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Zie ook
--------

[Kostenobjecten](cost-object.md)

[Kosteninvoer](cost-entries.md)

[Wat is nieuw of gewijzigd in Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)


