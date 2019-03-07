---
title: Serviceorders combineren
description: U kunt serviceorders combineren.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b94d81c431a068e891a0e05e996594f7e0be19f9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "311859"
---
# <a name="combine-service-orders"></a><span data-ttu-id="05596-103">Serviceorders combineren</span><span class="sxs-lookup"><span data-stu-id="05596-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="05596-104">Als u serviceorderregels automatisch maakt in het formulier **Serviceovereenkomsten**, kunt u een van de volgende opties kiezen om op te geven hoe u ze wilt groeperen:</span><span class="sxs-lookup"><span data-stu-id="05596-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="05596-105">**Per serviceovereenkomst**</span><span class="sxs-lookup"><span data-stu-id="05596-105">**By service agreement**</span></span>

  - <span data-ttu-id="05596-106">**Per servicetaak**</span><span class="sxs-lookup"><span data-stu-id="05596-106">**By service task**</span></span>

  - <span data-ttu-id="05596-107">**Per werknemer**</span><span class="sxs-lookup"><span data-stu-id="05596-107">**By employee**</span></span>

  - <span data-ttu-id="05596-108">**Per serviceobject**</span><span class="sxs-lookup"><span data-stu-id="05596-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="05596-109">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="05596-109">Example</span></span>

<span data-ttu-id="05596-110">U maakt een serviceovereenkomst waarvan de begindatum 31-03-2007 is.</span><span class="sxs-lookup"><span data-stu-id="05596-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="05596-111">In het veld **Serviceorders combineren** geeft u **Per serviceobject** op.</span><span class="sxs-lookup"><span data-stu-id="05596-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="05596-112">Vervolgens maakt u de volgende serviceovereenkomstregels:</span><span class="sxs-lookup"><span data-stu-id="05596-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05596-113">Overeenkomstregelnummer</span><span class="sxs-lookup"><span data-stu-id="05596-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="05596-114">Transactietype</span><span class="sxs-lookup"><span data-stu-id="05596-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="05596-115">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="05596-115">Description</span></span></p></th>
<th><p><span data-ttu-id="05596-116">Interval</span><span class="sxs-lookup"><span data-stu-id="05596-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="05596-117">Serviceobject</span><span class="sxs-lookup"><span data-stu-id="05596-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="05596-118">Begindatum</span><span class="sxs-lookup"><span data-stu-id="05596-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05596-119">1</span><span class="sxs-lookup"><span data-stu-id="05596-119">1</span></span></p></td>
<td><p><span data-ttu-id="05596-120"><strong>Uur</strong></span><span class="sxs-lookup"><span data-stu-id="05596-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="05596-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="05596-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="05596-122">Wekelijks</span><span class="sxs-lookup"><span data-stu-id="05596-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="05596-123">X-1</span><span class="sxs-lookup"><span data-stu-id="05596-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="05596-124">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="05596-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05596-125">2</span><span class="sxs-lookup"><span data-stu-id="05596-125">2</span></span></p></td>
<td><p><span data-ttu-id="05596-126"><strong>Uur</strong></span><span class="sxs-lookup"><span data-stu-id="05596-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="05596-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="05596-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="05596-128">Om de twee weken</span><span class="sxs-lookup"><span data-stu-id="05596-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="05596-129">X-2</span><span class="sxs-lookup"><span data-stu-id="05596-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="05596-130">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="05596-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05596-131">3</span><span class="sxs-lookup"><span data-stu-id="05596-131">3</span></span></p></td>
<td><p><span data-ttu-id="05596-132"><strong>Uur</strong></span><span class="sxs-lookup"><span data-stu-id="05596-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="05596-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="05596-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="05596-134">Wekelijks</span><span class="sxs-lookup"><span data-stu-id="05596-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="05596-135">X-2</span><span class="sxs-lookup"><span data-stu-id="05596-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="05596-136">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="05596-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="05596-137">U geeft geen tijdvensters voor de serviceovereenkomstregels op.</span><span class="sxs-lookup"><span data-stu-id="05596-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="05596-138">Daarom blijven de serviceorderregels staan op de datum waarop ze zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="05596-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="05596-139">Vervolgens genereert u vanuit het formulier **Serviceorders maken** serviceorderregels van 01-04-2007 tot 30-04-2007.</span><span class="sxs-lookup"><span data-stu-id="05596-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="05596-140">In totaal worden er tien serviceorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="05596-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="05596-141">Omdat u de door u geselecteerde gecombineerde instelling **Per serviceobject** is, krijgen alle serviceorders die worden gemaakt alleen serviceorderregels met één specifiek serviceobject.</span><span class="sxs-lookup"><span data-stu-id="05596-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="05596-142">Serviceorderregels die vanuit de serviceovereenkomst worden gegenereerd en dezelfde servicedatum en hetzelfde serviceobject hebben, worden gecombineerd tot één serviceorder.</span><span class="sxs-lookup"><span data-stu-id="05596-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="05596-143">In dit voorbeeld heeft de kalender die in het formulier <STRONG>Parameters voor servicebeheer</STRONG> is opgegeven, geen gesloten dagen.</span><span class="sxs-lookup"><span data-stu-id="05596-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="05596-144">Voor de aanvullende groepering van serviceorderregels tot serviceorders wordt uitgegaan van tijdvensters die u in de serviceovereenkomstregels opgeeft.</span><span class="sxs-lookup"><span data-stu-id="05596-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="05596-145">Zie ook</span><span class="sxs-lookup"><span data-stu-id="05596-145">See also</span></span>

[<span data-ttu-id="05596-146">Automatisch serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="05596-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


