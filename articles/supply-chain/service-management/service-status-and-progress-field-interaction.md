---
title: Interactie tussen servicestatuswaarden en het veld Voortgang
description: Het veld Voortgang in het formulier Serviceorders in de koptekst bevat de status van de gehele serviceorder, en de statusrapporten bevatten de status van de afzonderlijke regels van de serviceorder.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
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
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd70d00f7ce531b225362065dfd9f1f5c1adc754
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207319"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="b215e-103">Interactie tussen servicestatuswaarden en het veld Voortgang</span><span class="sxs-lookup"><span data-stu-id="b215e-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b215e-104">In het formulier **Serviceorders** bevat het veld **Voortgang** in de serviceorderkoptekst de status van de gehele serviceorder en bevatten de **status**rapporten de status van de afzonderlijke regels van de serviceorder.</span><span class="sxs-lookup"><span data-stu-id="b215e-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b215e-105">Voortgang</span><span class="sxs-lookup"><span data-stu-id="b215e-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="b215e-106">Status regel 1</span><span class="sxs-lookup"><span data-stu-id="b215e-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="b215e-107">Status regel 2</span><span class="sxs-lookup"><span data-stu-id="b215e-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="b215e-108">Status regel 3</span><span class="sxs-lookup"><span data-stu-id="b215e-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b215e-109"><strong>Onderhanden</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-110"><strong>Gemaakt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-111"><strong>Gemaakt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-112"><strong>Gemaakt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b215e-113"><strong>Onderhanden</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-114"><strong>Geannuleerd</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-115"><strong>Gemaakt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-116"><strong>Gemaakt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b215e-117"><strong>Onderhanden</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-118"><strong>Gemaakt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-119"><strong>Geannuleerd</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-120"><strong>Geboekt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b215e-121"><strong>Geannuleerd</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-122"><strong>Geannuleerd</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-123"><strong>Geannuleerd</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-124"><strong>Geannuleerd</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b215e-125"><strong>Geboekt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-126"><strong>Geboekt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-127"><strong>Geboekt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-128"><strong>Geboekt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b215e-129"><strong>Geboekt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-130"><strong>Geboekt</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-131"><strong>Geannuleerd</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b215e-132"><strong>Geannuleerd</strong></span><span class="sxs-lookup"><span data-stu-id="b215e-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b215e-133">De serviceorder is onderhanden als alle regels de status **Gemaakt** hebben en is nog steeds onderhanden als sommige regels de status **Geannuleerd** of **Geboekt** hebben.</span><span class="sxs-lookup"><span data-stu-id="b215e-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="b215e-134">Als alle regels in een serviceorder zijn gemarkeerd als **Geboekt**, is de voortgang van de statusorder **Geboekt**.</span><span class="sxs-lookup"><span data-stu-id="b215e-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="b215e-135">Als sommige regels de status **Geboekt** hebben terwijl andere regels de status **Geannuleerd** hebben, is de voortgangsstatus nog steeds **Geboekt**.</span><span class="sxs-lookup"><span data-stu-id="b215e-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


