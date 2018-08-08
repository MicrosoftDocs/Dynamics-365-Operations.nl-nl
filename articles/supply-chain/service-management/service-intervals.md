---
title: Service-intervallen
description: Met service-intervallen wordt aangegeven hoe vaak er serviceorderregels voor serviceovereenkomstregels worden gemaakt wanneer u serviceorders maakt.
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 10078cbd02209126e9655b823fcf844b692a4794
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="service-intervals"></a><span data-ttu-id="2c8f4-103">Service-intervallen</span><span class="sxs-lookup"><span data-stu-id="2c8f4-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c8f4-104">Met serviceovereenkomstintervallen wordt aangegeven hoe vaak er serviceorderregels voor serviceovereenkomstregels worden gemaakt wanneer u automatisch serviceorders maakt.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="2c8f4-105">Wanneer serviceorders automatisch worden gemaakt, worden serviceorderregels gemaakt vanaf de begindatum van de overeenkomstregel volgens het interval dat u voor de serviceovereenkomstregel hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="2c8f4-106">Als het veld **Interval** van een serviceovereenkomstregel op de pagina **Serviceovereenkomsten** leeg is, gaat het om een eenmalige gebeurtenis en wordt de regel niet gebruikt om steeds opnieuw serviceorders te maken.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="2c8f4-107">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2c8f4-107">Example</span></span>

<span data-ttu-id="2c8f4-108">Dit voorbeeld illustreert de invloed van een service-interval op serviceovereenkomstregels en die van serviceorderregels op een serviceorder.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="2c8f4-109">Een serviceovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="2c8f4-109">Create a service agreement</span></span>

<span data-ttu-id="2c8f4-110">U maakt eerst een serviceovereenkomst en stelt de optie **Serviceorders combineren** in op **Per serviceovereenkomst**.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="2c8f4-111">Klik op **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="2c8f4-112">Klik in het **actievenster** op het tabblad **Serviceovereenkomst** in de groep **Nieuw** op **Serviceovereenkomst** om een nieuwe serviceovereenkomst te maken.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="2c8f4-113">Voer een beschrijving in, selecteer een project in het veld **Project-id** en voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="2c8f4-114">In het veld **Serviceorders combineren** selecteert u **Per serviceovereenkomst**.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="2c8f4-115">U hebt nu de volgende serviceovereenkomst gemaakt:</span><span class="sxs-lookup"><span data-stu-id="2c8f4-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="2c8f4-116">Project</span><span class="sxs-lookup"><span data-stu-id="2c8f4-116">Project</span></span>      | <span data-ttu-id="2c8f4-117">Begindatum</span><span class="sxs-lookup"><span data-stu-id="2c8f4-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8f4-118">Uw project</span><span class="sxs-lookup"><span data-stu-id="2c8f4-118">Your project</span></span> | <span data-ttu-id="2c8f4-119">De datum die u voor het project hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-119">The date you specified for the project.</span></span> <span data-ttu-id="2c8f4-120">In dit voorbeeld wordt de huidige datum gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="2c8f4-121">Een serviceovereenkomstregel maken</span><span class="sxs-lookup"><span data-stu-id="2c8f4-121">Create a service agreement line</span></span>

<span data-ttu-id="2c8f4-122">Vervolgens maakt u een serviceovereenkomstregel die het transactietype **Uur** heeft.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="2c8f4-123">U voltooit dit deel van het voorbeeld door op de pagina **Service-intervallen** een service-interval van 10 dagen te maken.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="2c8f4-124">Selecteer de serviceovereenkomst die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="2c8f4-125">Ga naar het sneltabblad **Regels** en klik op de knop **Toevoegen** om een nieuwe regel te maken in het onderste deelvenster van de pagina **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="2c8f4-126">In het veld **Transactietype** selecteert u **Uur**.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="2c8f4-127">Selecteer in het veld **Werknemer** de werknemer die de service zal verzorgen.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="2c8f4-128">Selecteer het interval van 10 dagen in het veld **Service-interval**.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="2c8f4-129">U hebt nu een serviceovereenkomstregel gemaakt met de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="2c8f4-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="2c8f4-130">Transactietype</span><span class="sxs-lookup"><span data-stu-id="2c8f4-130">Transaction type</span></span> | <span data-ttu-id="2c8f4-131">Begindatum</span><span class="sxs-lookup"><span data-stu-id="2c8f4-131">Start date</span></span>                               | <span data-ttu-id="2c8f4-132">Dienstinterval</span><span class="sxs-lookup"><span data-stu-id="2c8f4-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="2c8f4-133">Uur</span><span class="sxs-lookup"><span data-stu-id="2c8f4-133">Hour</span></span>             | <span data-ttu-id="2c8f4-134">De huidige datum.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-134">The current date.</span></span>                        | <span data-ttu-id="2c8f4-135">Om de 10 dagen</span><span class="sxs-lookup"><span data-stu-id="2c8f4-135">Every 10 days</span></span>    |
| <span data-ttu-id="2c8f4-136">Werknemer</span><span class="sxs-lookup"><span data-stu-id="2c8f4-136">Worker</span></span>           | <span data-ttu-id="2c8f4-137">De werknemer die de service uitvoert.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="2c8f4-138">Er is geen tijdvenster voor de regel opgegeven.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="2c8f4-139">Geplande serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="2c8f4-139">Create planned service orders</span></span>

<span data-ttu-id="2c8f4-140">U kunt nu geplande serviceorders en serviceorderregels voor de volgende maand maken.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="2c8f4-141">Klik op de pagina **Serviceovereenkomsten** in het **actievenster** op het tabblad **Leveren** op **Geplande serviceorders**.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="2c8f4-142">Geef op de pagina **Serviceorders maken** de huidige datum in het veld **Begindatum** en een datum die één maand na de huidige datum ligt in het veld **Einddatum** op.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="2c8f4-143">Stel de schuifregelaar **Uur** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="2c8f4-144">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-144">Click **OK**.</span></span>

<span data-ttu-id="2c8f4-145">Omdat er geen groepering voor de serviceorder beschikbaar is (gedefinieerd via de optie **Per serviceovereenkomst** in het veld **Serviceorders combineren**), wordt voor elke serviceorder een serviceorderregel gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="2c8f4-146">Gemaakte serviceorders</span><span class="sxs-lookup"><span data-stu-id="2c8f4-146">Service orders created</span></span>

<span data-ttu-id="2c8f4-147">Er zijn drie serviceorderregels gemaakt binnen het tijdsbestek dat u hebt opgegeven in het dialoogvenster **Serviceorders maken**.</span><span class="sxs-lookup"><span data-stu-id="2c8f4-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="2c8f4-148">U kunt de serviceorderregels bekijken op de pagina **Serviceovereenkomsten** (**actievenster** \> **Leveren** (tabblad) \>**Weergeven** (knop).</span><span class="sxs-lookup"><span data-stu-id="2c8f4-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c8f4-149">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="2c8f4-149">Related topics</span></span>

[<span data-ttu-id="2c8f4-150">Service-intervallen instellen</span><span class="sxs-lookup"><span data-stu-id="2c8f4-150">Set up service intervals</span></span>](set-up-service-intervals.md)  


