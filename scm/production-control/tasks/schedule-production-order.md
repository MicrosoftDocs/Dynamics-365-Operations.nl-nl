--- 
title: Een productieorder plannen
description: Deze procedure toont hoe u een productieorder plant.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4aeb51fd2d9e916d5838b47c4a6b74800572a9ca
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="schedule-a-production-order"></a><span data-ttu-id="5cf6a-103">Een productieorder plannen</span><span class="sxs-lookup"><span data-stu-id="5cf6a-103">Schedule a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5cf6a-104">Deze procedure toont hoe u een productieorder plant.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="5cf6a-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5cf6a-106">Dit is de derde procedure van zeven die de productieorderlevenscyclus beschrijven.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="5cf6a-107">Een productieorder plannen</span><span class="sxs-lookup"><span data-stu-id="5cf6a-107">Schedule a production order</span></span>
1. <span data-ttu-id="5cf6a-108">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="5cf6a-109">Selecteer een productieorder met de status Geschat.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="5cf6a-110">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="5cf6a-111">Klik op Taken plannen.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="5cf6a-112">De parameters voor planning worden ingesteld op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="5cf6a-113">U kunt de parameters instellen voor specifieke gebruikers of alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="5cf6a-114">Selecteer in het veld Planningsrichting de optie 'Verder vanaf vandaag'.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="5cf6a-115">Voer in het veld Planningsdatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="5cf6a-116">Schakel het selectievakje Eindige capaciteit in of uit.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="5cf6a-117">Schakel het selectievakje Eindig materiaal in of uit.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="5cf6a-118">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="5cf6a-119">De resultaten van planning weergeven</span><span class="sxs-lookup"><span data-stu-id="5cf6a-119">View the scheduling results</span></span>
1. <span data-ttu-id="5cf6a-120">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="5cf6a-121">Klik op Alle taken.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-121">Click All jobs.</span></span>
    * <span data-ttu-id="5cf6a-122">Deze pagina toont de geplande taken die u zojuist hebt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="5cf6a-123">Vouw de sectie Planning uit of samen.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="5cf6a-124">Op het sneltabblad Planning kunt u de geplande datum en tijd weergeven.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="5cf6a-125">Klik op Query's.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-125">Click Inquiries.</span></span>
5. <span data-ttu-id="5cf6a-126">Klik op Capaciteitsbelasting.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-126">Click Capacity load.</span></span>
    * <span data-ttu-id="5cf6a-127">De pagina Capaciteitsbelasting toont de capaciteit die is gereserveerd via taakplanning, het totale aantal uren dat momenteel is gereserveerd voor de resource en het aantal uren dat beschikbaar is voor taakplanning voor de resource.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="5cf6a-128">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-128">Close the page.</span></span>
7. <span data-ttu-id="5cf6a-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-129">Close the page.</span></span>


