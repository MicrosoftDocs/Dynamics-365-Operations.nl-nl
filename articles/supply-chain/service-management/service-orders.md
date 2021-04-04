---
title: Serviceorders
description: Een serviceorder vertegenwoordigt het bezoek van een onderhoudsmonteur aan een klant op een bepaalde datum.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26a1c693be9581bd26ad43c70a024b0a8115afdf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254234"
---
# <a name="service-orders"></a><span data-ttu-id="b5224-103">Serviceorders</span><span class="sxs-lookup"><span data-stu-id="b5224-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b5224-104">Een serviceorder vertegenwoordigt het bezoek van een onderhoudsmonteur aan een klant op een bepaalde datum.</span><span class="sxs-lookup"><span data-stu-id="b5224-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="b5224-105">Elke serviceorder bestaat uit een of meer serviceorderregels.</span><span class="sxs-lookup"><span data-stu-id="b5224-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="b5224-106">Serviceorderregels vertegenwoordigen de uren werk die moeten worden uitgevoerd door de onderhoudsmonteur en de verwante artikelen, uitgaven en honoraria.</span><span class="sxs-lookup"><span data-stu-id="b5224-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="b5224-107">U kunt taken en objecten toevoegen aan een serviceorderregel.</span><span class="sxs-lookup"><span data-stu-id="b5224-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="b5224-108">U kunt vervolgens serviceorderregels groeperen volgens taak of object.</span><span class="sxs-lookup"><span data-stu-id="b5224-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="b5224-109">Ook kunt u artikelen uit de voorraad aan serviceorderregels koppelen.</span><span class="sxs-lookup"><span data-stu-id="b5224-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="b5224-110">Serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="b5224-110">Create service orders</span></span>

<span data-ttu-id="b5224-111">U kunt serviceorders maken aan de hand van serviceovereenkomsten en de regels voor die overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="b5224-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="b5224-112">U kunt echter alleen serviceorders maken die zijn gekoppeld aan een serviceovereenkomst tijdens de periode die is opgegeven in de overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="b5224-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="b5224-113">Als een serviceovereenkomst bijvoorbeeld geldig is voor het jaar 2011, kunt u serviceorders voor de overeenkomst maken van 1 januari 2011 en 31 December 2011.</span><span class="sxs-lookup"><span data-stu-id="b5224-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="b5224-114">U kunt ook serviceorders afzonderlijk maken, zonder deze te koppelen aan een overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="b5224-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="b5224-115">Deze serviceorders kunnen worden gebruikt om ongeplande of eenmalige onderhoudsbeurten te verwerken.</span><span class="sxs-lookup"><span data-stu-id="b5224-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="b5224-116">In maart wil een klant bijvoorbeeld behalve de machines die in de serviceovereenkomst staan opgegeven, nog twee andere machines laten onderhouden.</span><span class="sxs-lookup"><span data-stu-id="b5224-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="b5224-117">Voor deze taak maakt u serviceorders, maar u koppelt deze niet aan een overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="b5224-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b5224-118">Om serviceorders te maken die niet zijn gekoppeld aan een serviceovereenkomst, moet u het selectievakje <STRONG>Toestaan zonder serviceovereenkomst</STRONG> in het formulier <STRONG>Parameters voor servicebeheer</STRONG> aanvinken.</span><span class="sxs-lookup"><span data-stu-id="b5224-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="b5224-119">**Scenario's**</span><span class="sxs-lookup"><span data-stu-id="b5224-119">**Scenario**</span></span>

<span data-ttu-id="b5224-120">In het volgende scenario wordt een andere situatie beschreven waarin het handig een serviceorder te maken die niet is gekoppeld aan een serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="b5224-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="b5224-121">De verzender van het bedrijf ontvangt een oproep om noodonderhoud uit te voeren aan een lift.</span><span class="sxs-lookup"><span data-stu-id="b5224-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="b5224-122">Er is geen tijd om een serviceovereenkomst en een project voor de service in te stellen.</span><span class="sxs-lookup"><span data-stu-id="b5224-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="b5224-123">Daarom maakt de verzender een serviceorder rechtstreeks in het formulier **Serviceorders**, koppelt hij/zij de serviceorder aan een bestaand project en maakt hij/zij de serviceorderregels.</span><span class="sxs-lookup"><span data-stu-id="b5224-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="b5224-124">De verzender maakt ook een taak- of objectrelatie voor een bestaande serviceorder maken om het werk te registreren dat losstaat van de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="b5224-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="b5224-125">Zie voor meer informatie [Handmatig serviceorders maken](create-service-orders-manually.md) en [Servicetaakrelaties maken](create-service-task-relations.md).</span><span class="sxs-lookup"><span data-stu-id="b5224-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="b5224-126">De voortgang van serviceorders controleren</span><span class="sxs-lookup"><span data-stu-id="b5224-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="b5224-127">U kunt een fasesysteem en redencodes voor serviceorders instellen die een afspiegeling vormen van de voortgang van een serviceorder bij de diverse teams en werkzaamheden in het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="b5224-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="b5224-128">Voor elk stadium kunt u de acties opgeven die zijn toegestaan.</span><span class="sxs-lookup"><span data-stu-id="b5224-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="b5224-129">Zie voor meer informatie over redencodes [Redencodes maken](create-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b5224-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="b5224-130">**Voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="b5224-130">**Example**</span></span>

<span data-ttu-id="b5224-131">De verzender keurt een serviceorder goed.</span><span class="sxs-lookup"><span data-stu-id="b5224-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="b5224-132">De verzender werkt de fase van de serviceorder bij en geeft een redencode op die aangeeft dat de serviceorder is vrijgegeven aan de onderhoudsmonteur.</span><span class="sxs-lookup"><span data-stu-id="b5224-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="b5224-133">De onderhoudsmonteur gaat naar de klant en voert daar de werkzaamheden uit.</span><span class="sxs-lookup"><span data-stu-id="b5224-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="b5224-134">Artikelbehoeften voor serviceorders opgeven</span><span class="sxs-lookup"><span data-stu-id="b5224-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="b5224-135">U kunt de voorraadartikelen opgeven die vereist zijn voor serviceorders.</span><span class="sxs-lookup"><span data-stu-id="b5224-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="b5224-136">De serviceorder moet echter gekoppeld zijn aan een project.</span><span class="sxs-lookup"><span data-stu-id="b5224-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="b5224-137">Artikelbehoeften voor serviceorders worden verwerkt via een project.</span><span class="sxs-lookup"><span data-stu-id="b5224-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="b5224-138">**Voorbeeld**</span><span class="sxs-lookup"><span data-stu-id="b5224-138">**Example**</span></span>

<span data-ttu-id="b5224-139">De serviceorders die van de serviceovereenkomst zijn gemaakt, worden vervolgens verwerkt door de verzender.</span><span class="sxs-lookup"><span data-stu-id="b5224-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="b5224-140">Bij de eerste serviceorder realiseert de verzender zich dat de onderhoudsmonteur een belangrijk reserveonderdeel nodig heeft dat niet op voorraad is.</span><span class="sxs-lookup"><span data-stu-id="b5224-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="b5224-141">De verzender maakt rechtstreeks vanuit de serviceorder een artikelbehoefte voor het reserveonderdeel.</span><span class="sxs-lookup"><span data-stu-id="b5224-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="b5224-142">Regels verplaatsen en boeken</span><span class="sxs-lookup"><span data-stu-id="b5224-142">Move and post lines</span></span>

<span data-ttu-id="b5224-143">Een onderhoudsmonteur keert terug van een onderhoudsbeurt en wijzigt vervolgens de servicorderregels.</span><span class="sxs-lookup"><span data-stu-id="b5224-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="b5224-144">Tijdens het servicebezoek voerde de onderhoudsmonteur een onderhoudstaak uit die voor de volgende onderhoudsbeurt was gepland.</span><span class="sxs-lookup"><span data-stu-id="b5224-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="b5224-145">Daarom verplaatst de onderhoudsmonteur de regels van de volgende onderhoudsbeurt naar de huidige onderhoudsbeurt.</span><span class="sxs-lookup"><span data-stu-id="b5224-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="b5224-146">De onderhoudsmonteur boekt vervolgens de serviceorder.</span><span class="sxs-lookup"><span data-stu-id="b5224-146">The technician then posts the service order.</span></span> <span data-ttu-id="b5224-147">Zie voor meer informatie [Serviceorderregels verplaatsen](move-service-order-lines.md).</span><span class="sxs-lookup"><span data-stu-id="b5224-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="b5224-148">Serviceorders annuleren</span><span class="sxs-lookup"><span data-stu-id="b5224-148">Cancel service orders</span></span>

<span data-ttu-id="b5224-149">Een van de andere serviceorders die voor januari was gegenereerd, is vervallen omdat de taak is geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="b5224-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="b5224-150">De verzender annuleert daarom deze serviceorder.</span><span class="sxs-lookup"><span data-stu-id="b5224-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="b5224-151">Zie voor meer informatie [Serviceorders annuleren](cancel-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="b5224-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="b5224-152">Boeken vanuit projecten</span><span class="sxs-lookup"><span data-stu-id="b5224-152">Post from projects</span></span>

<span data-ttu-id="b5224-153">Aan het einde van elke week wil de verzender alle serviceorders van een bepaald project boeken.</span><span class="sxs-lookup"><span data-stu-id="b5224-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="b5224-154">Daarom zoekt de verzender het betreffende project in het formulier **Projecten** en boekt deze de serviceorders die zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="b5224-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="b5224-155">Zie voor meer informatie [Serviceorders boeken (klasseformulier)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="b5224-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="b5224-156">Serviceorders verwijderen</span><span class="sxs-lookup"><span data-stu-id="b5224-156">Delete service orders</span></span>

<span data-ttu-id="b5224-157">Tijdens de tweede helft van het jaar geeft de klant aan dat hij vaker een onderhoudsmonteur over de vloer wil hebben.</span><span class="sxs-lookup"><span data-stu-id="b5224-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="b5224-158">U moet een nieuwe, frequentere reeks onderhoudsbezoeken voor de resterende looptijd van de serviceovereenkomst maken.</span><span class="sxs-lookup"><span data-stu-id="b5224-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="b5224-159">U dient dus de reeds gemaakte serviceorders te verwijderen en nieuwe serviceorders te maken.</span><span class="sxs-lookup"><span data-stu-id="b5224-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="b5224-160">Zie voor meer informatie [Serviceorders verwijderen](delete-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="b5224-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b5224-161">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b5224-161">See also</span></span>

<span data-ttu-id="b5224-162">[Serviceorders (formulier)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="b5224-162">[Service orders (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]