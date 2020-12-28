---
title: Service-intervallen
description: Met service-intervallen wordt aangegeven hoe vaak er serviceorderregels voor serviceovereenkomstregels worden gemaakt wanneer u serviceorders maakt.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1027a6a1ddb1057ba039382d394522d6f9538a90
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425531"
---
# <a name="service-intervals"></a><span data-ttu-id="811cb-103">Service-intervallen</span><span class="sxs-lookup"><span data-stu-id="811cb-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="811cb-104">Met serviceovereenkomstintervallen wordt aangegeven hoe vaak er serviceorderregels voor serviceovereenkomstregels worden gemaakt wanneer u automatisch serviceorders maakt.</span><span class="sxs-lookup"><span data-stu-id="811cb-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="811cb-105">Wanneer serviceorders automatisch worden gemaakt, worden serviceorderregels gemaakt vanaf de begindatum van de overeenkomstregel volgens het interval dat u voor de serviceovereenkomstregel hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="811cb-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="811cb-106">Als het veld **Interval** van een serviceovereenkomstregel op de pagina **Serviceovereenkomsten** leeg is, gaat het om een eenmalige gebeurtenis en wordt de regel niet gebruikt om steeds opnieuw serviceorders te maken.</span><span class="sxs-lookup"><span data-stu-id="811cb-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="811cb-107">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="811cb-107">Example</span></span>

<span data-ttu-id="811cb-108">Dit voorbeeld illustreert de invloed van een service-interval op serviceovereenkomstregels en die van serviceorderregels op een serviceorder.</span><span class="sxs-lookup"><span data-stu-id="811cb-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="811cb-109">Een serviceovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="811cb-109">Create a service agreement</span></span>

<span data-ttu-id="811cb-110">U maakt eerst een serviceovereenkomst en stelt de optie **Serviceorders combineren** in op **Per serviceovereenkomst**.</span><span class="sxs-lookup"><span data-stu-id="811cb-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="811cb-111">Klik op **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="811cb-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="811cb-112">Klik in het **actievenster** op het tabblad **Serviceovereenkomst** in de groep **Nieuw** op **Serviceovereenkomst** om een nieuwe serviceovereenkomst te maken.</span><span class="sxs-lookup"><span data-stu-id="811cb-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="811cb-113">Voer een beschrijving in, selecteer een project in het veld **Project-id** en voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="811cb-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="811cb-114">In het veld **Serviceorders combineren** selecteert u **Per serviceovereenkomst**.</span><span class="sxs-lookup"><span data-stu-id="811cb-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="811cb-115">U hebt nu de volgende serviceovereenkomst gemaakt:</span><span class="sxs-lookup"><span data-stu-id="811cb-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="811cb-116">Project</span><span class="sxs-lookup"><span data-stu-id="811cb-116">Project</span></span>      | <span data-ttu-id="811cb-117">Begindatum</span><span class="sxs-lookup"><span data-stu-id="811cb-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="811cb-118">Uw project</span><span class="sxs-lookup"><span data-stu-id="811cb-118">Your project</span></span> | <span data-ttu-id="811cb-119">De datum die u voor het project hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="811cb-119">The date you specified for the project.</span></span> <span data-ttu-id="811cb-120">In dit voorbeeld wordt de huidige datum gebruikt.</span><span class="sxs-lookup"><span data-stu-id="811cb-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="811cb-121">Een serviceovereenkomstregel maken</span><span class="sxs-lookup"><span data-stu-id="811cb-121">Create a service agreement line</span></span>

<span data-ttu-id="811cb-122">Vervolgens maakt u een serviceovereenkomstregel die het transactietype **Uur** heeft.</span><span class="sxs-lookup"><span data-stu-id="811cb-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="811cb-123">U voltooit dit deel van het voorbeeld door op de pagina **Service-intervallen** een service-interval van 10 dagen te maken.</span><span class="sxs-lookup"><span data-stu-id="811cb-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="811cb-124">Selecteer de serviceovereenkomst die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="811cb-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="811cb-125">Ga naar het sneltabblad **Regels** en klik op de knop **Toevoegen** om een nieuwe regel te maken in het onderste deelvenster van de pagina **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="811cb-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="811cb-126">In het veld **Transactietype** selecteert u **Uur**.</span><span class="sxs-lookup"><span data-stu-id="811cb-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="811cb-127">Selecteer in het veld **Werknemer** de werknemer die de service zal verzorgen.</span><span class="sxs-lookup"><span data-stu-id="811cb-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="811cb-128">Selecteer het interval van 10 dagen in het veld **Service-interval**.</span><span class="sxs-lookup"><span data-stu-id="811cb-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="811cb-129">U hebt nu een serviceovereenkomstregel gemaakt met de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="811cb-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="811cb-130">Transactietype</span><span class="sxs-lookup"><span data-stu-id="811cb-130">Transaction type</span></span> | <span data-ttu-id="811cb-131">Begindatum</span><span class="sxs-lookup"><span data-stu-id="811cb-131">Start date</span></span>                               | <span data-ttu-id="811cb-132">Dienstinterval</span><span class="sxs-lookup"><span data-stu-id="811cb-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="811cb-133">Uur</span><span class="sxs-lookup"><span data-stu-id="811cb-133">Hour</span></span>             | <span data-ttu-id="811cb-134">De huidige datum.</span><span class="sxs-lookup"><span data-stu-id="811cb-134">The current date.</span></span>                        | <span data-ttu-id="811cb-135">Om de 10 dagen</span><span class="sxs-lookup"><span data-stu-id="811cb-135">Every 10 days</span></span>    |
| <span data-ttu-id="811cb-136">Werknemer</span><span class="sxs-lookup"><span data-stu-id="811cb-136">Worker</span></span>           | <span data-ttu-id="811cb-137">De werknemer die de service uitvoert.</span><span class="sxs-lookup"><span data-stu-id="811cb-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="811cb-138">Er is geen tijdvenster voor de regel opgegeven.</span><span class="sxs-lookup"><span data-stu-id="811cb-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="811cb-139">Geplande serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="811cb-139">Create planned service orders</span></span>

<span data-ttu-id="811cb-140">U kunt nu geplande serviceorders en serviceorderregels voor de volgende maand maken.</span><span class="sxs-lookup"><span data-stu-id="811cb-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="811cb-141">Klik op de pagina **Serviceovereenkomsten** in het **actievenster** op het tabblad **Leveren** op **Geplande serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="811cb-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="811cb-142">Geef op de pagina **Serviceorders maken** de huidige datum in het veld **Begindatum** en een datum die één maand na de huidige datum ligt in het veld **Einddatum** op.</span><span class="sxs-lookup"><span data-stu-id="811cb-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="811cb-143">Stel de schuifregelaar **Uur** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="811cb-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="811cb-144">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="811cb-144">Click **OK**.</span></span>

<span data-ttu-id="811cb-145">Omdat er geen groepering voor de serviceorder beschikbaar is (gedefinieerd via de optie **Per serviceovereenkomst** in het veld **Serviceorders combineren**), wordt voor elke serviceorder een serviceorderregel gemaakt.</span><span class="sxs-lookup"><span data-stu-id="811cb-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="811cb-146">Gemaakte serviceorders</span><span class="sxs-lookup"><span data-stu-id="811cb-146">Service orders created</span></span>

<span data-ttu-id="811cb-147">Er zijn drie serviceorderregels gemaakt binnen het tijdsbestek dat u hebt opgegeven in het dialoogvenster **Serviceorders maken**.</span><span class="sxs-lookup"><span data-stu-id="811cb-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="811cb-148">U kunt de serviceorderregels bekijken op de pagina **Serviceovereenkomsten** (**actievenster** \> **Leveren** (tabblad) \>**Weergeven** (knop)).</span><span class="sxs-lookup"><span data-stu-id="811cb-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="811cb-149">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="811cb-149">Related topics</span></span>

[<span data-ttu-id="811cb-150">Service-intervallen instellen</span><span class="sxs-lookup"><span data-stu-id="811cb-150">Set up service intervals</span></span>](set-up-service-intervals.md)  

