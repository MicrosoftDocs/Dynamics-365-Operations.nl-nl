---
title: Ondersteuning van kanbanoverboekingsbord voor streepjescodescanners
description: Het kanbanoverboekingsbord ondersteunt scannerinvoer vanuit een widgetstreepjescodescanner om een kanbantaak te selecteren, starten, voltooien en legen.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aedfe7ef96d62401b1d0de0f2cd035036c68e51a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007061"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a>Ondersteuning van kanbanoverboekingsbord voor streepjescodescanners

[!include [banner](../includes/banner.md)]

Het kanbanoverboekingsbord ondersteunt scannerinvoer vanuit een widgetstreepjescodescanner om een kanbantaak te selecteren, starten, voltooien en legen.

<a name="registration-modes"></a>Registratiemodi
------------------

Op het sneltabblad **Scannerregistratie** kunt u de registratiemodus selecteren die de actie bepaalt bij het scannen van een kanbankaartnummer of het handmatig invoeren van het nummer in het veld Kanbankaartnummer.

| Registratiemodus instellen | Beschrijving                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| Beginnen                 | Registreert een kanbanoverboekingstaak als in uitvoering.                                                 |
| Voltooid              | Registreert een kanbanoverboekingstaak als voltooid.                                                   |
| Leeg                 | Registreert de materiaalverwerkingseenheid waarnaar door een kanbankaart wordt verwezen als leeg.              |
| Selecteren                | Registreert een kanbankaartnummer en selecteert automatisch de taak waarnaar wordt verwezen in de kanbanlijst. |

 
<a name="registration-mode-select"></a>Registratiemodus Selecteren
------------------------

Wanneer u een streepjescodelezer gebruikt om een taak te selecteren, wordt de weergavemodus van het kanbanbord gewijzigd. In deze modus gelden de volgende voorwaarden:

-   Alleen de gescande kanbantaak wordt weergegeven.
-   De details van de geselecteerde taak worden weergegeven op het sneltabblad **Details**.
-   Het sneltabblad **Berichten** geeft alleen berichten weer voor de geselecteerde taak.
-   U kunt de status van de taak wijzigen met de functies die beschikbaar zijn in het Actievenster. Het kanbanoverboekingsbord blijft één taak weergeven tijdens deze periode.
-   U kunt de gegevens in de lijst met taken handmatig bijwerken door te klikken op **Vernieuwen** (Shift+F5) in het actievenster. Nadat u de gegevens hebt vernieuwd, worden de volledige resultaten voor het taakfilter opnieuw weergegeven.

## <a name="job-status-and-possible-actions"></a>Taakstatus en mogelijke acties
De status van de geselecteerde taak en de status van alle getraceerde taken voor gebeurteniskanbans bepalen of u de taak verder kunt verwerken. De volgende tabel bevat informatie over deze statussen en taken:
-   De statussen die beschikbaar zijn voor taken of voor de materiaalverwerkingseenheden waarnaar wordt verwezen door de taken.
-   Elke taak die u voor de taak kunt uitvoeren.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th>Functietype</th>
<th>Taakstatus of de status van materiaalverwerkingseenheid</th>
<th>Orderverzamellijst bijwerken</th>
<th>Beginnen</th>
<th>Registratie bijwerken</th>
<th>Voltooid</th>
<th>Leeg</th>
<th>Gebeurteniskanbans maken</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Overboeken</td>
<td><ul>
<li>Niet gepland</li>
<li>Er zijn geen getraceerde taken of getraceerde taken zijn Voltooid</li>
</ul></td>
<td>Ja</td>
<td>Ja</td>
<td>Ja</td>
<td>Ja</td>
<td>Nee</td>
<td>Ja</td>
</tr>
<tr class="even">
<td>Overboeken</td>
<td><ul>
<li>Niet gepland</li>
<li>De getraceerde taak is niet Voltooid</li>
</ul></td>
<td>Ja</td>
<td>Nee</td>
<td>Ja</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
</tr>
<tr class="odd">
<td>Overboeken</td>
<td>In uitvoering</td>
<td>Ja</td>
<td>Nee</td>
<td>Ja</td>
<td>Ja</td>
<td>Nee</td>
<td>Nee</td>
</tr>
<tr class="even">
<td>Overboeken</td>
<td>Voltooid</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Ja</td>
<td>Nee</td>
</tr>
<tr class="odd">
<td>Overboeken of verwerken</td>
<td>Leeg</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
</tr>
<tr class="even">
<td>Overboeken of verwerken</td>
<td>Er is geen kanbankaart gevonden</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
</tr>
<tr class="odd">
<td>Overboeken of verwerken</td>
<td>Er is een kanbankaart gevonden, maar deze is niet toegewezen aan een kanban</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
</tr>
<tr class="even">
<td>Verwerken</td>
<td><ul>
<li>Niet gepland</li>
<li>Voorbereid</li>
<li>In uitvoering</li>
</ul></td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
</tr>
<tr class="odd">
<td>Verwerken</td>
<td>Voltooid</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
<td>Nee</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]