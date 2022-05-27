---
title: Interactie tussen servicestatuswaarden en het veld Voortgang
description: Het veld Voortgang in het formulier Serviceorders in de koptekst bevat de status van de gehele serviceorder, en de statusrapporten bevatten de status van de afzonderlijke regels van de serviceorder.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e83df9ca8ee19b5e29d4eccf2bd883ee6ddff62
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677641"
---
# <a name="service-status-and-progress-field-interaction"></a>Interactie tussen servicestatuswaarden en het veld Voortgang

[!include [banner](../includes/banner.md)]

In het formulier **Serviceorders** bevat het veld **Voortgang** in de serviceorderkoptekst de status van de gehele serviceorder en bevatten de **status** rapporten de status van de afzonderlijke regels van de serviceorder.

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Voortgang</p></th>
<th><p>Status regel 1</p></th>
<th><p>Status regel 2</p></th>
<th><p>Status regel 3</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Onderhanden</strong></p></td>
<td><p><strong>Gemaakt</strong></p></td>
<td><p><strong>Gemaakt</strong></p></td>
<td><p><strong>Gemaakt</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Onderhanden</strong></p></td>
<td><p><strong>Geannuleerd</strong></p></td>
<td><p><strong>Gemaakt</strong></p></td>
<td><p><strong>Gemaakt</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Onderhanden</strong></p></td>
<td><p><strong>Gemaakt</strong></p></td>
<td><p><strong>Geannuleerd</strong></p></td>
<td><p><strong>Geboekt</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Geannuleerd</strong></p></td>
<td><p><strong>Geannuleerd</strong></p></td>
<td><p><strong>Geannuleerd</strong></p></td>
<td><p><strong>Geannuleerd</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Geboekt</strong></p></td>
<td><p><strong>Geboekt</strong></p></td>
<td><p><strong>Geboekt</strong></p></td>
<td><p><strong>Geboekt</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Geboekt</strong></p></td>
<td><p><strong>Geboekt</strong></p></td>
<td><p><strong>Geannuleerd</strong></p></td>
<td><p><strong>Geannuleerd</strong></p></td>
</tr>
</tbody>
</table>

De serviceorder is onderhanden als alle regels de status **Gemaakt** hebben en is nog steeds onderhanden als sommige regels de status **Geannuleerd** of **Geboekt** hebben.

Als alle regels in een serviceorder zijn gemarkeerd als **Geboekt**, is de voortgang van de statusorder **Geboekt**. Als sommige regels de status **Geboekt** hebben terwijl andere regels de status **Geannuleerd** hebben, is de voortgangsstatus nog steeds **Geboekt**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
